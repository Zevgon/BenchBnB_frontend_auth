{
  current_user: {
    id: 1,
    username: "biff"
  },
  languages: {
    1: {
      id: 2,
      name: 'German',
    },
    2: {
      id: 4,
      name: 'Italian'
    }
  },
  nodes: {
    1: {
      id: 6,
      languageId: 2
      completed: false,
      unlocked: true
      words: {
        1: {
          nodeId: 6,
          word: 'ein',
          translation: ['one', 'a', 'an'],
          answeredCorrectly; false
        },
        2: {
          nodeId: 6,
          word: 'ich',
          translation: ['I'],
          answeredCorrectly: true
        },
        3: etc.
      }
    },
    2: etc.
  },
  forms: {
    signUp: {
      errors: ['password too short']
    },
    signIn: {
      errors: []
    }
  }
}
